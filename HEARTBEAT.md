## PeopleOS Check-in

**时间窗口：** 仅在 13:00–23:00 执行，超出范围 → `HEARTBEAT_OK`

### 选人逻辑

扫描所有 `./peopleos/*/` 目录，找到每个 person 最新的日期文件（`YYYY-MM-DD.md`）：

**先过滤：** 该 person 最新的记录文件在过去 18 小时内有过写入（文件修改时间）→ 跳过，关系还热着，不需要介入。

**再排优先级（从剩余候选中选一个）：**

1. 有超过 2 天未跟进的 `[action]`，且 `[stance]` 条目密度高
2. 有超过 3 天未跟进的 `[action]`
3. 最近 2 天内有新 `[fact]` 但没有后续，且 `[stance]` 条目密度高
4. 最近 3 天内有新 `[fact]` 但没有后续
5. 超过 5 天没有任何新条目，且 `[stance]` 条目密度高
6. 超过 7 天没有任何新条目

没有任何候选 → `HEARTBEAT_OK`

读取 `./peopleos/heartbeat-state.json`，跳过 `lastPersonAsked` 中记录的上一个人（防止用户忽略消息时重复问同一个人）。

### 发送内容

合并成一条消息自然发出，不分条列举。以具体的人/事切入，末尾留软开口。

**没有 person 目录时：** 发一次：
> "最近怎么样，有没有什么在心里搁着的？"

之后每次 heartbeat 检查：`./peopleos/` 下仍无 person 目录 → `HEARTBEAT_OK`，不重复发送。

### 发送后

更新 `./peopleos/heartbeat-state.json`：
```json
{
  "lastPersonAsked": "<person 名字，无 person 时为 null>",
  "lastAskedAt": "<ISO 时间戳>"
}
```
