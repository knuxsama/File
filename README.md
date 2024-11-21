## Student Login
### Request
```json
{
  "username": String,
  "teacher_unique_code": Int,
}
```

### Response Success
```json
{
  "status_code": Int,
  "message": String,
  "data": {
    "username": String,
    "teacher_unique_code": Int
  }
}
```

### Response Failed
```json
{
  "status_code": Int,
  "message": String,
  "data": null
}
```

## Student Get Exam (Per BAB)
### Request
```json
{
  "chapter_id": Int
  "teacher_unique_code": Int,
}
```

### Response Success
```json
{
  "status_code": Int,
  "message": String,
  "data": {
    "all_question": [
      {
        "uid": String,
        "question": String,
        "number": Int,
        "answer": Array<String>,
        "picture": String,
        "correct_answer": String
      },
      ...
    ]
  }
}
```

### Response Failed
```json
{
  "status_code": Int,
  "message": String,
  "data": null
}
```

## Student Submit Exam (Per BAB)
### Request
```json
{
  "chapter_id": Int
  "username": String,
  "score": Int
}
```

### Response Success
```json
{
  "status_code": Int,
  "message": String,
}
```

### Response Failed
```json
{
  "status_code": Int,
  "message": String,
}
```

## Teacher Get All Student Score
### Request
```json
{
  "chapter_id": Int,
  "teacher_unique_code": Int,
}
```

### Response Success
```json
{
  "status_code": Int,
  "message": String,
  "data": [
    {
      "student_username": String,
      "score": Int
    },
    ...
  ]
}
```

### Response Failed
```json
{
  "status_code": Int,
  "message": String,
  "data": null
}
```
