<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فيديو الولاية - ضاغط الفيديو الاحترافي</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #6C63FF;
            --primary-light: #a29cff;
            --secondary-color: #FF6584;
            --dark-color: #2D3748;
            --light-color: #F7FAFC;
            --gray-color: #E2E8F0;
            --success-color: #48BB78;
            --warning-color: #ED8936;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Tajawal', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            color: var(--dark-color);
            line-height: 1.6;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px 0;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary-color);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .logo-icon {
            margin-left: 10px;
            font-size: 2.8rem;
        }
        
        .subtitle {
            color: var(--dark-color);
            font-size: 1.2rem;
            opacity: 0.8;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .app-container {
            background-color: white;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            padding: 40px;
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
        }
        
        .app-container::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
        }
        
        .upload-section {
            text-align: center;
            padding: 60px 20px;
            border: 2px dashed var(--gray-color);
            border-radius: 12px;
            margin-bottom: 40px;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            background-color: var(--light-color);
        }
        
        .upload-section:hover {
            border-color: var(--primary-color);
            background-color: rgba(108, 99, 255, 0.05);
            transform: translateY(-3px);
        }
        
        .upload-icon {
            font-size: 60px;
            color: var(--primary-color);
            margin-bottom: 20px;
            transition: all 0.3s;
        }
        
        .upload-section:hover .upload-icon {
            transform: scale(1.1);
        }
        
        .upload-text h2 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--dark-color);
        }
        
        .upload-text p {
            color: #718096;
            font-size: 1rem;
        }
        
        .file-input {
            display: none;
        }
        
        .settings {
            margin-bottom: 40px;
        }
        
        .settings-header {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }
        
        .settings-icon {
            font-size: 1.8rem;
            color: var(--primary-color);
            margin-left: 15px;
        }
        
        .settings h2 {
            color: var(--dark-color);
            font-size: 1.5rem;
            margin-bottom: 0;
        }
        
        .settings-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        label {
            display: block;
            margin-bottom: 12px;
            font-weight: 600;
            color: var(--dark-color);
            font-size: 1.1rem;
        }
        
        select {
            width: 100%;
            padding: 14px 18px;
            border: 1px solid var(--gray-color);
            border-radius: 10px;
            background-color: white;
            font-size: 1rem;
            color: var(--dark-color);
            appearance: none;
            background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='currentColor' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3e%3cpolyline points='6 9 12 15 18 9'%3e%3c/polyline%3e%3c/svg%3e");
            background-repeat: no-repeat;
            background-position: right 15px center;
            background-size: 1em;
            transition: all 0.3s;
        }
        
        select:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(108, 99, 255, 0.2);
            outline: none;
        }
        
        .range-container {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.03);
            border: 1px solid var(--gray-color);
        }
        
        input[type="range"] {
            -webkit-appearance: none;
            width: 100%;
            height: 10px;
            background: var(--gray-color);
            border-radius: 5px;
            margin-top: 15px;
            margin-bottom: 25px;
            transition: all 0.3s;
        }
        
        input[type="range"]:hover {
            background: #cbd5e0;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 24px;
            height: 24px;
            background: var(--primary-color);
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 2px 6px rgba(108, 99, 255, 0.4);
            transition: all 0.3s;
        }
        
        input[type="range"]::-webkit-slider-thumb:hover {
            transform: scale(1.1);
            box-shadow: 0 4px 8px rgba(108, 99, 255, 0.5);
        }
        
        .range-labels {
            display: flex;
            justify-content: space-between;
            margin-top: 5px;
        }
        
        .range-label {
            font-size: 0.9rem;
            color: #718096;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .range-label.active {
            color: var(--primary-color);
            font-weight: 600;
        }
        
        .range-label i {
            font-size: 1.2rem;
            margin-bottom: 5px;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            background-color: var(--primary-color);
            color: white;
            padding: 16px 32px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s;
            box-shadow: 0 4px 6px rgba(108, 99, 255, 0.2);
        }
        
        .btn:hover {
            background-color: var(--primary-light);
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(108, 99, 255, 0.3);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .btn i {
            margin-left: 8px;
            font-size: 1.2rem;
        }
        
        .btn-secondary {
            background-color: white;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
            box-shadow: none;
        }
        
        .btn-secondary:hover {
            background-color: rgba(108, 99, 255, 0.05);
            color: var(--primary-light);
            border-color: var(--primary-light);
        }
        
        .btn-disabled {
            background-color: #CBD5E0;
            cursor: not-allowed;
            box-shadow: none;
        }
        
        .btn-disabled:hover {
            transform: none;
            background-color: #CBD5E0;
        }
        
        .action-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }
        
        .progress-container {
            display: none;
            margin-top: 40px;
            text-align: center;
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }
        
        .progress-title {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: var(--dark-color);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .progress-title i {
            margin-left: 10px;
            color: var(--primary-color);
            font-size: 1.5rem;
        }
        
        .progress-bar {
            width: 100%;
            height: 12px;
            background-color: var(--gray-color);
            border-radius: 6px;
            margin-bottom: 15px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            width: 0%;
            transition: width 0.4s ease;
            border-radius: 6px;
        }
        
        .progress-text {
            font-size: 1rem;
            color: #718096;
        }
        
        .result-section {
            display: none;
            margin-top: 40px;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .result-header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .result-header h2 {
            font-size: 1.8rem;
            color: var(--dark-color);
            margin-bottom: 10px;
        }
        
        .result-header p {
            color: #718096;
            font-size: 1.1rem;
        }
        
        .video-preview {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .video-container {
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
        }
        
        .video-container:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }
        
        .video-container h3 {
            margin-bottom: 20px;
            color: var(--dark-color);
            font-size: 1.3rem;
            display: flex;
            align-items: center;
        }
        
        .video-container h3 i {
            margin-left: 10px;
            color: var(--primary-color);
        }
        
        video {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            background-color: #000;
        }
        
        .file-info {
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
            font-size: 0.95rem;
            color: #718096;
        }
        
        .file-info span {
            display: flex;
            align-items: center;
        }
        
        .file-info i {
            margin-left: 5px;
        }
        
        .stats {
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            margin-top: 30px;
        }
        
        .stats-title {
            font-size: 1.3rem;
            color: var(--dark-color);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
        }
        
        .stats-title i {
            margin-left: 10px;
            color: var(--primary-color);
        }
        
        .stat-item {
            display: flex;
            justify-content: space-between;
            padding: 15px 0;
            border-bottom: 1px solid var(--gray-color);
            align-items: center;
        }
        
        .stat-item:last-child {
            border-bottom: none;
        }
        
        .stat-label {
            display: flex;
            align-items: center;
            font-size: 1.1rem;
        }
        
        .stat-label i {
            margin-left: 10px;
            color: #718096;
        }
        
        .stat-value {
            font-weight: 700;
            font-size: 1.1rem;
        }
        
        .success {
            color: var(--success-color);
        }
        
        .warning {
            color: var(--warning-color);
        }
        
        .result-actions {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }
        
        @media (max-width: 768px) {
            .app-container {
                padding: 25px;
            }
            
            .video-preview {
                grid-template-columns: 1fr;
            }
            
            .action-buttons, .result-actions {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <span>فيديو الولاية</span>
                <i class="fas fa-video logo-icon"></i>
            </div>
            <p class="subtitle">أداة ضغط الفيديو الاحترافية - قلل حجم ملفاتك مع الحفاظ على الجودة العالية</p>
        </header>
        
        <div class="app-container">
            <div class="upload-section" id="uploadArea">
                <div class="upload-icon">
                    <i class="fas fa-cloud-upload-alt"></i>
                </div>
                <div class="upload-text">
                    <h2>اسحب وأسقط ملف الفيديو هنا</h2>
                    <p>أو انقر لاختيار ملف (يدعم MP4, MOV, AVI, MKV بحد أقصى 2GB)</p>
                </div>
                <input type="file" id="fileInput" class="file-input" accept="video/*">
            </div>
            
            <div class="settings">
                <div class="settings-header">
                    <i class="fas fa-sliders-h settings-icon"></i>
                    <h2>إعدادات الضغط</h2>
                </div>
                
                <div class="settings-grid">
                    <div class="form-group">
                        <label for="compressionLevel"><i class="fas fa-compress-alt"></i> مستوى الضغط</label>
                        <div class="range-container">
                            <input type="range" id="compressionLevel" min="0" max="100" value="50">
                            <div class="range-labels">
                                <div class="range-label" data-value="0">
                                    <i class="fas fa-star"></i>
                                    <span>جودة عالية</span>
                                </div>
                                <div class="range-label active" data-value="50">
                                    <i class="fas fa-balance-scale"></i>
                                    <span>متوازن</span>
                                </div>
                                <div class="range-label" data-value="100">
                                    <i class="fas fa-weight-hanging"></i>
                                    <span>حجم صغير</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="outputFormat"><i class="fas fa-file-video"></i> تنسيق المخرجات</label>
                        <select id="outputFormat">
                            <option value="mp4">MP4 (موصى به)</option>
                            <option value="webm">WebM</option>
                            <option value="mov">MOV</option>
                            <option value="avi">AVI</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="resolution"><i class="fas fa-expand"></i> الدقة</label>
                        <select id="resolution">
                            <option value="original">الأصلية</option>
                            <option value="2160">4K (2160p)</option>
                            <option value="1080">1080p (Full HD)</option>
                            <option value="720">720p (HD)</option>
                            <option value="480">480p (SD)</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="quality"><i class="fas fa-crown"></i> جودة الفيديو</label>
                        <select id="quality">
                            <option value="high">عالية (موصى به)</option>
                            <option value="medium">متوسطة</option>
                            <option value="low">منخفضة</option>
                        </select>
                    </div>
                </div>
            </div>
            
            <div class="action-buttons">
                <button id="compressBtn" class="btn btn-disabled" disabled>
                    <i class="fas fa-compress-arrows-alt"></i> اضغط الفيديو
                </button>
                <button id="resetBtn" class="btn btn-secondary" disabled>
                    <i class="fas fa-redo"></i> إعادة تعيين
                </button>
            </div>
            
            <div class="progress-container" id="progressContainer">
                <div class="progress-title">
                    <i class="fas fa-spinner fa-spin"></i>
                    <span>جاري ضغط الفيديو...</span>
                </div>
                <div class="progress-bar">
                    <div class="progress" id="progressBar"></div>
                </div>
                <p class="progress-text" id="progressText">0% مكتمل</p>
            </div>
            
            <div class="result-section" id="resultSection">
                <div class="result-header">
                    <h2>تم ضغط الفيديو بنجاح!</h2>
                    <p>يمكنك الآن معاينة النتائج وتحميل الفيديو المضغوط</p>
                </div>
                
                <div class="video-preview">
                    <div class="video-container">
                        <h3>
                            <i class="fas fa-file-video"></i>
                            <span>الفيديو الأصلي</span>
                        </h3>
                        <video controls id="originalVideo"></video>
                        <div class="file-info">
                          
