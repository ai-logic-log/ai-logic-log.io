import React, { useState, useEffect, useMemo } from 'react';
import { 
  History, 
  PlusCircle, 
  Calendar as CalendarIcon, 
  TrendingUp, 
  ClipboardList, 
  Lock, 
  ChevronLeft, 
  ChevronRight, 
  User, 
  Trash2, 
  Clock, 
  Search, 
  BarChart3, 
  AlertCircle,
  Info,
  Zap,
  MessageSquareQuote,
  BrainCircuit,
  ShieldCheck
} from 'lucide-react';

// --- 전역 설정 ---
const PROFESSOR_PASSWORD = "2026";
const STORAGE_KEY = "ai_logic_log_data_2026";

export default function App() {
  const [view, setView] = useState('home'); 
  const [logs, setLogs] = useState([]);
  const [role, setRole] = useState('student');
  const [isProfAuth, setIsProfAuth] = useState(false);
  const [passInput, setPassInput] = useState("");
  const [loading, setLoading] = useState(false);

  const [formData, setFormData] = useState({
    studentName: '',
    studentId: '',
    assignmentTitle: '', 
    step: 'idea', 
    aiTool: '', 
    prompt: '', 
    criticalReflection: '', 
    logDate: new Date().toISOString().split('T')[0]
  });

  // 1. 데이터 불러오기 (Local Storage)
  useEffect(() => {
    const savedData = localStorage.getItem(STORAGE_KEY);
    if (savedData) {
      try {
        setLogs(JSON.parse(savedData));
      } catch (e) {
        console.error("데이터 로드 실패", e);
      }
    }
  }, []);

  // 2. 데이터 저장
  const saveLog = (e) => {
    e.preventDefault();
    setLoading(true);
    
    const newLog = {
      ...formData,
      id: Date.now().toString(),
      createdAt: new Date().toISOString()
    };

    const updatedLogs = [newLog, ...logs];
    setLogs(updatedLogs);
    localStorage.setItem(STORAGE_KEY, JSON.stringify(updatedLogs));
    
    setTimeout(() => {
      setLoading(false);
      alert("성공적으로 기록되었습니다.");
      setView('myLogs');
    }, 500);
  };

  // 3. 데이터 삭제
  const deleteLog = (id) => {
    if (window.confirm("이 기록을 삭제하시겠습니까?")) {
      const updatedLogs = logs.filter(log => log.id !== id);
      setLogs(updatedLogs);
      localStorage.setItem(STORAGE_KEY, JSON.stringify(updatedLogs));
    }
  };

  const handleRoleChange = (newRole) => {
    setRole(newRole);
    setIsProfAuth(false);
    setView('home');
  };

  const verifyProfessor = (e) => {
    e.preventDefault();
    if (passInput === PROFESSOR_PASSWORD) {
      setIsProfAuth(true);
      setView('dashboard');
    } else {
      alert("암호가 일치하지 않습니다.");
    }
  };

  return (
    <div className="min-h-screen bg-[#F8FAFF] text-slate-900 font-sans selection:bg-indigo-100">
      {/* Navigation */}
      <nav className="bg-white border-b border-slate-100 sticky top-0 z-40 shadow-sm backdrop-blur-md bg-white/80">
        <div className="max-w-6xl mx-auto px-6 h-16 flex items-center justify-between">
          <div className="flex items-center gap-2 cursor-pointer group" onClick={() => setView('home')}>
            <div className="bg-indigo-600 p-2 rounded-xl text-white group-hover:rotate-12 transition-transform">
              <History className="w-5 h-5" />
            </div>
            <span className="font-bold text-xl tracking-tighter text-indigo-950">AI LogicLog <span className="text-xs font-normal text-slate-300 ml-1 italic">v2.2 (GitHub)</span></span>
          </div>
          
          <div className="flex items-center gap-2 sm:gap-4">
            {role === 'student' && (
              <button onClick={() => setView('myLogs')} className={`flex items-center gap-2 px-3 py-2 rounded-xl text-sm font-bold transition ${view === 'myLogs' ? 'bg-indigo-50 text-indigo-700' : 'text-slate-500 hover:bg-slate-50'}`}>
                <TrendingUp className="w-4 h-4" /> 내 성장 기록
              </button>
            )}
            <button onClick={() => setView('calendar')} className={`flex items-center gap-2 px-3 py-2 rounded-xl text-sm font-bold transition ${view === 'calendar' ? 'bg-indigo-50 text-indigo-700' : 'text-slate-500 hover:bg-slate-50'}`}>
              <CalendarIcon className="w-4 h-4" /> 기록 달력
            </button>
            <select 
              value={role} 
              onChange={(e) => handleRoleChange(e.target.value)}
              className="bg-slate-50 border-none rounded-xl px-3 py-2 text-xs font-bold focus:ring-2 focus:ring-indigo-500 outline-none cursor-pointer"
            >
              <option value="student">학생 모드</option>
              <option value="professor">교수자 모드</option>
            </select>
          </div>
        </div>
      </nav>

      <main className="max-w-6xl mx-auto px-6 py-8">
        {role === 'professor' && !isProfAuth ? (
          <div className="max-w-md mx-auto mt-20 p-10 bg-white rounded-[2.5rem] shadow-2xl border border-slate-100 text-center space-y-8 animate-in zoom-in-95 duration-500">
            <div className="bg-indigo-50 w-20 h-20 rounded-full flex items-center justify-center mx-auto text-indigo-600">
              <Lock className="w-10 h-10" />
            </div>
            <div className="space-y-2">
              <h2 className="text-3xl font-black tracking-tight text-slate-900">교수자 인증</h2>
              <p className="text-slate-500 text-sm leading-relaxed">전체 사고 과정을 검토하려면 암호를 입력하세요.</p>
            </div>
            <form onSubmit={verifyProfessor} className="space-y-4">
              <input 
                type="password" value={passInput} onChange={e => setPassInput(e.target.value)}
                placeholder="Password"
                className="w-full px-6 py-4 rounded-2xl border border-slate-200 focus:ring-4 focus:ring-indigo-500/10 outline-none text-center text-2xl tracking-[0.5em]"
              />
              <div className="p-4 bg-amber-50 rounded-2xl border border-amber-100 flex items-center gap-3">
                <Info className="w-5 h-5 text-amber-600 shrink-0" />
                <div className="text-left">
                  <span className="text-[10px] text-amber-600 uppercase font-black block mb-0.5">Admin Key Hint</span>
                  <span className="text-xl font-black text-indigo-600">{PROFESSOR_PASSWORD}</span>
                </div>
              </div>
              <button type="submit" className="w-full py-4 bg-indigo-600 text-white rounded-2xl font-bold text-lg hover:bg-indigo-700 transition shadow-xl shadow-indigo-100 active:scale-[0.98]">
                대시보드 접속
              </button>
            </form>
          </div>
        ) : (
          <div className="animate-in fade-in duration-500">
            {view === 'home' && <HomeView role={role} setView={setView} />}
            {view === 'log' && <LogFormView formData={formData} setFormData={setFormData} onSave={saveLog} loading={loading} setView={setView} />}
            {view === 'dashboard' && <ProfessorDashboard logs={logs} deleteLog={deleteLog} />}
            {view === 'calendar' && <CalendarView logs={logs} />}
            {view === 'myLogs' && <StudentGrowthView logs={logs} defaultInfo={{ name: formData.studentName, id: formData.studentId }} />}
          </div>
        )}
      </main>
    </div>
  );
}

// --- 하위 뷰 컴포넌트들 ---

function HomeView({ role, setView }) {
  return (
    <div className="py-20 text-center space-y-12 max-w-4xl mx-auto">
      <div className="space-y-6">
        <div className="inline-block px-4 py-1.5 bg-indigo-50 text-indigo-600 rounded-full text-xs font-black tracking-widest uppercase">
          AI Ethics & Critical Thinking Portfolio
        </div>
        <h1 className="text-6xl font-black text-slate-900 tracking-tight leading-[1.1]">
          AI를 활용하는 당신의 <br /><span className="text-indigo-600">논리적 궤적</span>을 남기세요
        </h1>
        <p className="text-xl text-slate-500 leading-relaxed font-medium">
          저장된 데이터는 브라우저에 안전하게 보관되며,<br />
          당신의 비판적 성찰 기록은 훌륭한 학습 포트폴리오가 됩니다.
        </p>
      </div>
      
      <div className="flex flex-wrap justify-center gap-4">
        {role === 'student' ? (
          <>
            <button onClick={() => setView('log')} className="bg-indigo-600 text-white px-10 py-5 rounded-[2rem] font-bold text-xl hover:bg-indigo-700 shadow-2xl shadow-indigo-100 flex items-center gap-3 transition-all hover:scale-105 active:scale-95">
              <PlusCircle className="w-6 h-6" /> 새 로그 기록하기
            </button>
            <button onClick={() => setView('myLogs')} className="bg-white border-2 border-slate-100 text-slate-700 px-10 py-5 rounded-[2rem] font-bold text-xl hover:bg-slate-50 shadow-sm flex items-center gap-3 transition-all hover:scale-105 active:scale-95">
              <TrendingUp className="w-6 h-6 text-indigo-600" /> 내 타임라인 보기
            </button>
          </>
        ) : (
          <button onClick={() => setView('dashboard')} className="bg-slate-900 text-white px-12 py-5 rounded-[2rem] font-bold text-xl hover:bg-black shadow-2xl shadow-slate-200 flex items-center gap-3 transition-all hover:scale-105 active:scale-95">
            <ClipboardList className="w-6 h-6" /> 전체 과정 모니터링
          </button>
        )}
      </div>

      <div className="grid md:grid-cols-3 gap-8 text-left pt-16">
        <FeatureCard icon={<MessageSquareQuote className="text-indigo-600" />} title="질문 기록" desc="AI에게 입력한 프롬프트를 보관하여 질문의 발전 과정을 추적합니다." />
        <FeatureCard icon={<Zap className="text-amber-500" />} title="비판적 성찰" desc="AI 답변 중 어떤 오류를 찾았고 어떻게 수정했는지 명시합니다." />
        <FeatureCard icon={<BarChart3 className="text-emerald-500" />} title="데이터 보존" desc="Firebase 없이 LocalStorage를 사용하여 독립적으로 작동합니다." />
      </div>
    </div>
  );
}

function LogFormView({ formData, setFormData, onSave, loading, setView }) {
  const STEPS = [
    { id: 'idea', label: '아이디어' },
    { id: 'outline', label: '개요작성' },
    { id: 'draft', label: '초안작성' },
    { id: 'fact-check', label: '사실확인' },
    { id: 'editing', label: '최종편집' }
  ];

  return (
    <div className="max-w-4xl mx-auto bg-white rounded-[2.5rem] shadow-2xl shadow-indigo-100/50 border border-slate-100 overflow-hidden">
      <div className="bg-indigo-600 p-10 text-white relative">
        <h2 className="text-4xl font-black tracking-tight">AI Interaction Log</h2>
        <p className="text-indigo-100 mt-2 text-lg font-medium">작성하신 내용은 현재 브라우저의 저장소에 기록됩니다.</p>
        <BrainCircuit className="absolute -right-10 -top-10 w-64 h-64 text-white opacity-10 rotate-12" />
      </div>

      <form onSubmit={onSave} className="p-10 space-y-10">
        <div className="grid md:grid-cols-2 gap-8 bg-slate-50/50 p-8 rounded-[2rem] border border-slate-100 shadow-inner">
          <InputGroup label="작성자 성함" value={formData.studentName} onChange={v => setFormData({...formData, studentName: v})} placeholder="성함 입력" />
          <InputGroup label="학번" value={formData.studentId} onChange={v => setFormData({...formData, studentId: v})} placeholder="학번 입력" />
        </div>

        <div className="space-y-8">
          <div className="grid md:grid-cols-2 gap-8">
            <div className="space-y-6">
              <InputGroup label="과제 제목" value={formData.assignmentTitle} onChange={v => setFormData({...formData, assignmentTitle: v})} placeholder="진행 중인 과제명" />
              <div>
                <label className="block text-sm font-black text-slate-700 mb-3 ml-1 uppercase">진행 단계</label>
                <div className="grid grid-cols-5 gap-2">
                  {STEPS.map(s => (
                    <button 
                      key={s.id} type="button" onClick={() => setFormData({...formData, step: s.id})}
                      className={`py-2 rounded-xl text-[10px] font-black border transition ${formData.step === s.id ? 'bg-indigo-600 text-white border-indigo-600 shadow-lg' : 'bg-white text-slate-400 border-slate-200 hover:border-indigo-300'}`}
                    >
                      {s.label}
                    </button>
                  ))}
                </div>
              </div>
              <div className="flex gap-4">
                <InputGroup label="사용 AI" value={formData.aiTool} onChange={v => setFormData({...formData, aiTool: v})} placeholder="ChatGPT 등" flex />
                <InputGroup label="날짜" type="date" value={formData.logDate} onChange={v => setFormData({...formData, logDate: v})} flex />
              </div>
            </div>

            <div className="space-y-6">
              <div>
                <label className="block text-sm font-black text-slate-700 mb-2 ml-1 uppercase">입력 프롬프트</label>
                <textarea 
                  required rows="5" value={formData.prompt}
                  onChange={e => setFormData({...formData, prompt: e.target.value})}
                  className="w-full px-5 py-4 rounded-2xl border border-slate-200 focus:ring-4 focus:ring-indigo-500/10 outline-none transition resize-none text-sm"
                  placeholder="AI에게 무엇을 질문했나요?"
                />
              </div>
              <div>
                <label className="block text-sm font-black text-indigo-600 mb-2 ml-1 flex items-center gap-1 uppercase">
                  <Zap className="w-4 h-4" /> 비판적 성찰 및 재구성
                </label>
                <textarea 
                  required rows="5" value={formData.criticalReflection}
                  onChange={e => setFormData({...formData, criticalReflection: e.target.value})}
                  className="w-full px-5 py-4 rounded-2xl border-2 border-indigo-100 bg-indigo-50/20 focus:ring-4 focus:ring-indigo-500/10 outline-none transition resize-none text-sm"
                  placeholder="AI의 답변 중 보완하거나 수정한 내용은 무엇인가요?"
                />
              </div>
            </div>
          </div>
        </div>

        <div className="flex gap-4 pt-6">
          <button type="button" onClick={() => setView('home')} className="flex-1 py-5 text-slate-400 font-bold hover:text-slate-600">취소</button>
          <button type="submit" disabled={loading} className="flex-[3] py-5 bg-indigo-600 text-white rounded-2xl font-bold text-xl hover:bg-indigo-700 shadow-xl transition-all active:scale-[0.98]">
            {loading ? "저장 중..." : "로컬 저장소에 기록 저장"}
          </button>
        </div>
      </form>
    </div>
  );
}

function StudentGrowthView({ logs, defaultInfo }) {
  const [searchName, setSearchName] = useState(defaultInfo.name || "");
  const [searchId, setSearchId] = useState(defaultInfo.id || "");
  const [isSearched, setIsSearched] = useState(!!(defaultInfo.name && defaultInfo.id));

  const myLogs = useMemo(() => {
    if (!searchName || !searchId) return [];
    return logs.filter(l => l.studentName === searchName && l.studentId === searchId)
               .sort((a, b) => new Date(a.logDate) - new Date(b.logDate));
  }, [logs, searchName, searchId]);

  return (
    <div className="space-y-10 max-w-5xl mx-auto">
      <div className="bg-white p-8 rounded-[2rem] border border-slate-200 shadow-sm flex flex-col md:flex-row gap-6 items-center justify-between">
        <div>
          <h2 className="text-3xl font-black text-slate-900 tracking-tight">나의 성장 타임라인</h2>
          <p className="text-slate-500 mt-1 font-medium italic">브라우저에 기록된 당신의 사유를 확인하세요.</p>
        </div>
        <div className="flex gap-2 w-full md:w-auto">
          <input type="text" value={searchName} onChange={e => setSearchName(e.target.value)} placeholder="이름" className="flex-1 md:w-32 px-4 py-3 rounded-xl border border-slate-200 text-sm" />
          <input type="text" value={searchId} onChange={e => setSearchId(e.target.value)} placeholder="학번" className="flex-1 md:w-40 px-4 py-3 rounded-xl border border-slate-200 text-sm" />
          <button onClick={() => setIsSearched(true)} className="bg-indigo-600 text-white px-6 py-3 rounded-xl font-bold active:scale-95"><Search className="w-5 h-5" /></button>
        </div>
      </div>

      {!isSearched ? (
        <div className="py-20 text-center text-slate-300">
          <History className="w-20 h-20 mx-auto mb-6 opacity-20" />
          <p className="text-lg font-medium">정보를 입력하여 기록을 조회하세요.</p>
        </div>
      ) : myLogs.length === 0 ? (
        <div className="py-20 text-center bg-white rounded-[2rem] border border-dashed border-slate-200">
          <AlertCircle className="w-16 h-16 mx-auto mb-4 text-slate-200" />
          <p className="text-slate-500 font-medium">해당 정보로 조회된 기록이 없습니다.</p>
        </div>
      ) : (
        <div className="space-y-8 relative">
          <div className="absolute left-6 top-0 bottom-0 w-1 bg-indigo-50 hidden sm:block" />
          {myLogs.map((log, idx) => (
            <div key={log.id} className="relative pl-0 sm:pl-16 group">
              <div className="absolute left-[18px] top-2 w-4 h-4 rounded-full bg-indigo-600 border-4 border-white shadow-md z-10 hidden sm:block" />
              <div className="bg-white p-8 rounded-[2.5rem] border border-slate-200 shadow-sm hover:shadow-lg transition-all">
                <div className="flex justify-between items-start mb-6">
                  <div>
                    <span className="text-[10px] font-black uppercase bg-indigo-50 text-indigo-600 px-3 py-1 rounded-lg">{log.step}</span>
                    <h4 className="text-2xl font-black text-slate-900 mt-2">{log.assignmentTitle}</h4>
                  </div>
                  <div className="text-xs font-bold text-slate-400 bg-slate-50 px-3 py-1.5 rounded-full">{log.logDate}</div>
                </div>
                <div className="space-y-4">
                  <div className="bg-slate-50 p-4 rounded-xl italic text-sm text-slate-600 shadow-inner">"{log.prompt}"</div>
                  <div className="bg-indigo-50/50 p-5 rounded-xl text-sm text-slate-800 border border-indigo-100">{log.criticalReflection}</div>
                </div>
              </div>
            </div>
          ))}
        </div>
      )}
    </div>
  );
}

function CalendarView({ logs }) {
  const [current, setCurrent] = useState(new Date());
  const [selectedLogs, setSelectedLogs] = useState([]);
  const [selectedStr, setSelectedStr] = useState("");

  const daysInMonth = new Date(current.getFullYear(), current.getMonth() + 1, 0).getDate();
  const startDay = new Date(current.getFullYear(), current.getMonth(), 1).getDay();
  const label = current.toLocaleString('ko-KR', { month: 'long', year: 'numeric' });

  const onClickDay = (day) => {
    const d = new Date(current.getFullYear(), current.getMonth(), day).toISOString().split('T')[0];
    const found = logs.filter(l => l.logDate === d);
    setSelectedLogs(found);
    setSelectedStr(d);
  };

  return (
    <div className="grid lg:grid-cols-5 gap-8">
      <div className="lg:col-span-3 bg-white rounded-[2.5rem] shadow-sm border border-slate-200 p-10">
        <div className="flex items-center justify-between mb-10">
          <h2 className="text-3xl font-black text-slate-900">{label}</h2>
          <div className="flex gap-2">
            <button onClick={() => setCurrent(new Date(current.getFullYear(), current.getMonth() - 1))} className="p-3 hover:bg-slate-50 rounded-2xl"><ChevronLeft /></button>
            <button onClick={() => setCurrent(new Date(current.getFullYear(), current.getMonth() + 1))} className="p-3 hover:bg-slate-50 rounded-2xl"><ChevronRight /></button>
          </div>
        </div>
        <div className="grid grid-cols-7 gap-4">
          {['일','월','화','수','목','금','토'].map(d => <div key={d} className="text-center text-[10px] font-black text-slate-400 uppercase tracking-widest mb-4">{d}</div>)}
          {Array.from({length: startDay}).map((_, i) => <div key={`e-${i}`} />)}
          {Array.from({length: daysInMonth}).map((_, i) => {
            const day = i + 1;
            const targetDate = new Date(current.getFullYear(), current.getMonth(), day).toISOString().split('T')[0];
            const count = logs.filter(l => l.logDate === targetDate).length;
            return (
              <button 
                key={day} onClick={() => onClickDay(day)}
                className={`h-20 rounded-3xl flex flex-col items-center justify-center border-2 transition-all ${count > 0 ? 'bg-indigo-50 border-indigo-200 shadow-sm' : 'bg-slate-50/50 border-transparent text-slate-300'}`}
              >
                <span className="text-lg font-black">{day}</span>
                {count > 0 && <span className="text-[10px] font-bold text-indigo-600 mt-1">{count} Logs</span>}
              </button>
            );
          })}
        </div>
      </div>
      <div className="lg:col-span-2">
        <div className="bg-slate-900 text-white rounded-[2.5rem] p-10 h-full shadow-2xl relative overflow-hidden min-h-[500px]">
          <Clock className="absolute -right-6 -bottom-6 w-48 h-48 opacity-5" />
          <h3 className="text-2xl font-bold mb-8 flex items-center gap-3">{selectedStr || '날짜를 선택하세요'}</h3>
          <div className="space-y-4">
            {selectedLogs.length === 0 ? (
              <div className="text-center py-20 opacity-30">기록이 없습니다.</div>
            ) : (
              selectedLogs.map(log => (
                <div key={log.id} className="bg-white/5 border border-white/10 p-6 rounded-3xl">
                  <div className="flex justify-between items-center mb-2">
                    <span className="text-[10px] font-black bg-indigo-500/20 text-indigo-300 px-3 py-1 rounded-full uppercase">{log.step}</span>
                    <span className="text-[10px] text-slate-500 font-bold">{log.studentName}</span>
                  </div>
                  <h4 className="font-bold text-lg">{log.assignmentTitle}</h4>
                </div>
              ))
            )}
          </div>
        </div>
      </div>
    </div>
  );
}

function ProfessorDashboard({ logs, deleteLog }) {
  const grouped = useMemo(() => {
    const res = {};
    logs.forEach(l => {
      const key = `${l.studentName} (${l.studentId})`;
      if (!res[key]) res[key] = [];
      res[key].push(l);
    });
    return Object.entries(res);
  }, [logs]);

  return (
    <div className="space-y-10">
      <header className="flex justify-between items-center">
        <div>
          <h2 className="text-4xl font-black text-slate-900 tracking-tight">전체 사고 모니터링</h2>
          <p className="text-slate-500 mt-1 font-medium">수집된 로컬 로그 데이터 (Total: {logs.length})</p>
        </div>
        <div className="bg-indigo-600 text-white px-5 py-2.5 rounded-2xl text-sm font-black flex items-center gap-2 shadow-lg shadow-indigo-100">
          <ShieldCheck className="w-5 h-5" /> Admin Verified
        </div>
      </header>

      <div className="grid gap-10">
        {grouped.length === 0 ? (
          <div className="py-40 text-center bg-white rounded-[3rem] border border-slate-100">
            <ClipboardList className="w-20 h-20 mx-auto mb-4 opacity-10" />
            <p className="text-slate-400 font-medium">저장된 데이터가 없습니다.</p>
          </div>
        ) : (
          grouped.map(([student, sLogs]) => (
            <div key={student} className="bg-white rounded-[3rem] border border-slate-200 overflow-hidden shadow-sm">
              <div className="bg-slate-50 p-8 border-b border-slate-200 flex justify-between items-center">
                <div className="flex items-center gap-4">
                  <div className="bg-white p-3 rounded-2xl border border-slate-200"><User className="w-6 h-6 text-indigo-600" /></div>
                  <h3 className="font-black text-xl text-slate-800">{student}</h3>
                </div>
              </div>
              <div className="p-8 overflow-x-auto">
                <table className="w-full text-left text-sm min-w-[800px]">
                  <thead>
                    <tr className="text-slate-400 text-[10px] uppercase tracking-widest border-b border-slate-100">
                      <th className="pb-6 pl-4">날짜/단계</th>
                      <th className="pb-6 w-1/4">과제</th>
                      <th className="pb-6 w-1/4">프롬프트</th>
                      <th className="pb-6 w-1/4 text-indigo-600">성찰(Reflection)</th>
                      <th className="pb-6 text-center pr-4">제어</th>
                    </tr>
                  </thead>
                  <tbody className="divide-y divide-slate-50">
                    {sLogs.map(log => (
                      <tr key={log.id} className="hover:bg-slate-50/50 transition-colors">
                        <td className="py-6 pl-4">
                          <div className="font-black">{log.logDate}</div>
                          <div className="text-[10px] text-indigo-600 font-black uppercase">{log.step}</div>
                        </td>
                        <td className="py-6">
                          <div className="font-bold text-slate-700">{log.assignmentTitle}</div>
                          <div className="text-[10px] text-slate-400 font-bold">{log.aiTool}</div>
                        </td>
                        <td className="py-6 pr-6">
                          <div className="text-xs text-slate-500 italic line-clamp-2 bg-slate-50 p-2 rounded-lg">"{log.prompt}"</div>
                        </td>
                        <td className="py-6 pr-6">
                          <div className="text-xs font-semibold text-slate-800 bg-indigo-50/30 p-4 rounded-2xl border border-indigo-100/30">{log.criticalReflection}</div>
                        </td>
                        <td className="py-6 text-center pr-4">
                          <button onClick={() => deleteLog(log.id)} className="text-slate-200 hover:text-red-500 p-2"><Trash2 className="w-5 h-5" /></button>
                        </td>
                      </tr>
                    ))}
                  </tbody>
                </table>
              </div>
            </div>
          ))
        )}
      </div>
    </div>
  );
}

function FeatureCard({ icon, title, desc }) {
  return (
    <div className="bg-white p-10 rounded-[2.5rem] border border-slate-100 shadow-sm hover:shadow-xl transition-all">
      <div className="bg-slate-50 w-16 h-16 rounded-[1.5rem] flex items-center justify-center mb-6 text-3xl shadow-inner">{icon}</div>
      <h3 className="font-black text-2xl mb-3 tracking-tight text-slate-900">{title}</h3>
      <p className="text-slate-500 leading-relaxed text-sm font-medium">{desc}</p>
    </div>
  );
}

function InputGroup({ label, value, onChange, placeholder, type="text", flex }) {
  return (
    <div className={flex ? 'flex-1' : 'w-full'}>
      <label className="block text-xs font-black text-slate-400 uppercase tracking-widest mb-3 ml-1">{label}</label>
      <input 
        type={type} required value={value}
        onChange={e => onChange(e.target.value)}
        placeholder={placeholder}
        className="w-full px-6 py-4 rounded-2xl border border-slate-200 focus:ring-4 focus:ring-indigo-500/10 outline-none transition font-semibold text-slate-700 shadow-sm"
      />
    </div>
  );
}
