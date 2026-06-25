# TABLES:

1. Users:
    id
    full_name
    email
    password
    role
    profile_picture
    created_at
    updated_at

2. Documents:
    id
    user_id
    title
    original_filename
    stored_filename
    file_type
    file_size
    upload_date
    status

3. Summaries:
    id
    document_id
    summary_text
    generated_at

4. Flashcards:
    id
    document_id
    question
    answer
    difficulty

5. Quiz:
    id
    document_id
    title
    total_questions
    created_at

6. Questions:
    id
    quiz_id
    question
    option_a
    option_b
    option_c
    option_d
    correct_answer
    explanation
    difficulty

7. Chat History:
    id
    user_id
    document_id
    question
    answer
    created_at

8. Progress:
    id
    user_id
    documents_read
    quiz_attempted
    average_score
    study_time
    last_active

9. Study Session:
    id
    user_id
    start_time
    end_time
    duration

10. AI Request: [IMP]
    id
    user_id
    request_type
    tokens_used
    processing_time
    status
    created_at