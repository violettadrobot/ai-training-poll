import React, { useState } from 'react';
import { TrendingUp, DollarSign, Clock, AlertCircle, Linkedin, Mail } from 'lucide-react';

export default function ModernROICalculator() {
  const [trainingCost, setTrainingCost] = useState(5000);
  const [employeeCount, setEmployeeCount] = useState(1);
  const [salaryType, setSalaryType] = useState('average');
  const [averageSalary, setAverageSalary] = useState(100000);
  const [employees, setEmployees] = useState([{ salary: 100000 }]);
  const [activities, setActivities] = useState([
    { name: 'Email Triage', hoursSavedPerDay: 2 },
    { name: 'Benefits Q&A', hoursSavedPerDay: 1 },
    { name: 'Onboarding', hoursSavedPerDay: 0.5 }
  ]);
  const [activeTab, setActiveTab] = useState('overview');
  const [workDaysPerYear] = useState(250);

  const handleEmployeeCountChange = (e) => {
    const count = parseInt(e.target.value) || 1;
    setEmployeeCount(count);
    const newEmployees = Array(count).fill(null).map((_, i) => ({
      salary: employees[i]?.salary || averageSalary
    }));
    setEmployees(newEmployees);
  };

  const handleEmployeeSalaryChange = (index, value) => {
    const newEmployees = [...employees];
    newEmployees[index].salary = parseFloat(value) || 0;
    setEmployees(newEmployees);
  };

  const handleActivityChange = (index, field, value) => {
    const newActivities = [...activities];
    newActivities[index][field] = field === 'name' ? value : parseFloat(value) || 0;
    setActivities(newActivities);
  };

  const addActivity = () => {
    setActivities([...activities, { name: '', hoursSavedPerDay: 0 }]);
  };

  const removeActivity = (index) => {
    setActivities(activities.filter((_, i) => i !== index));
  };

  const calculateSalaries = () => {
    if (salaryType === 'average') {
      return Array(employeeCount).fill(averageSalary);
    }
    return employees.map(e => e.salary);
  };

  const calculateHourlyRate = (salary) => salary / 2080;

  const calculateTotalHoursSaved = () => {
    return activities.reduce((total, activity) => {
      return total + (activity.hoursSavedPerDay * workDaysPerYear);
    }, 0);
  };

  const calculateBenefit = () => {
    const salaries = calculateSalaries();
    let totalBenefit = 0;

    activities.forEach(activity => {
      const hoursSaved = activity.hoursSavedPerDay * workDaysPerYear;
      salaries.forEach(salary => {
        const hourlyRate = calculateHourlyRate(salary);
        totalBenefit += hoursSaved * hourlyRate;
      });
    });

    return totalBenefit;
  };

  const totalBenefit = calculateBenefit();
  const netBenefit = totalBenefit - trainingCost;
  const roi = trainingCost > 0 ? ((totalBenefit - trainingCost) / trainingCost * 100).toFixed(0) : 0;
  const monthlyBenefit = totalBenefit / 12;
  const breakEvenMonths = (trainingCost / monthlyBenefit).toFixed(2);
  const breakEvenDays = Math.round(breakEvenMonths * 30);
  const totalHoursSaved = calculateTotalHoursSaved();
  const averageHourlyRate = calculateSalaries().reduce((a, b) => a + b, 0) / employeeCount / 2080;
  const costPerHour = trainingCost / totalHoursSaved;

  const BreakEvenTimeline = () => {
    const months = [1, 3, 6, 12];
    return (
      <div className="space-y-4">
        <div className="grid grid-cols-4 gap-2">
          {months.map((month) => {
            const cumBenefit = monthlyBenefit * month;
            const cumProfit = cumBenefit - trainingCost;
            const isBreakEven = month >= Math.ceil(breakEvenMonths);
            return (
              <div key={month} className={`p-3 rounded-lg border-2 transition-all ${isBreakEven ? 'border-[#06B6D4] bg-[#0C4F64]' : 'border-[#334155] bg-[#1E293B]'}`}>
                <p className="text-xs font-semibold mb-1" style={{ color: '#F1F5F9' }}>Month {month}</p>
                <p className={`text-sm font-bold ${isBreakEven ? '' : ''}`} style={{ color: isBreakEven ? '#FCD34D' : '#F1F5F9' }}>
                  ${cumProfit.toLocaleString('en-US', { maximumFractionDigits: 0 })}
                </p>
                <p className="text-xs mt-1 font-medium" style={{ color: '#F1F5F9' }}>{isBreakEven ? '✓ Positive' : `${(Math.ceil(breakEvenMonths) - month)} mo to BE`}</p>
              </div>
            );
          })}
        </div>
      </div>
    );
  };

  return (
    <div className="w-full min-h-screen" style={{ backgroundColor: '#0F172A' }}>
      {/* Header */}
      <div className="border-b" style={{ borderColor: '#1E293B', backgroundColor: '#0F172A' }}>
        <div className="max-w-7xl mx-auto px-6 py-12">
          <div className="flex items-center gap-3 mb-3">
            <div className="w-1 h-8" style={{ backgroundColor: '#06B6D4' }}></div>
            <h1 className="text-4xl font-bold" style={{ color: '#F1F5F9' }}>AI Training ROI Calculator</h1>
          </div>
          <p style={{ color: '#CBD5E1' }}>Calculate the financial impact of AI training on your HR team</p>
        </div>
      </div>

      {/* Tab Navigation */}
      <div className="border-b" style={{ borderColor: '#1E293B', backgroundColor: '#0F172A' }}>
        <div className="max-w-7xl mx-auto px-6 flex gap-4">
          <button
            onClick={() => setActiveTab('overview')}
            className={`px-6 py-4 font-medium transition-all border-b-2 ${activeTab === 'overview' ? 'border-[#06B6D4]' : 'border-transparent'}`}
            style={{ color: activeTab === 'overview' ? '#06B6D4' : '#CBD5E1' }}
          >
            Calculator
          </button>
          <button
            onClick={() => setActiveTab('breakeven')}
            className={`px-6 py-4 font-medium transition-all border-b-2 ${activeTab === 'breakeven' ? 'border-[#06B6D4]' : 'border-transparent'}`}
            style={{ color: activeTab === 'breakeven' ? '#06B6D4' : '#CBD5E1' }}
          >
            Break-Even Analysis
          </button>
        </div>
      </div>

      <div className="max-w-7xl mx-auto px-6 py-8">
        {/* CALCULATOR TAB - SPLIT LAYOUT */}
        {activeTab === 'overview' && (
          <div className="grid grid-cols-2 gap-8">
            {/* LEFT SIDE - INPUTS */}
            <div className="space-y-6">
              {/* Training Cost */}
              <div className="p-6 rounded-lg" style={{ backgroundColor: '#1E293B' }}>
                <h3 className="text-lg font-bold mb-4" style={{ color: '#F1F5F9' }}>Training Investment</h3>
                <div>
                  <label className="block text-sm mb-2" style={{ color: '#CBD5E1' }}>Training Cost ($)</label>
                  <input
                    type="number"
                    value={trainingCost}
                    onChange={(e) => setTrainingCost(parseFloat(e.target.value) || 0)}
                    className="w-full px-4 py-3 rounded-lg border-2 text-white"
                    style={{ backgroundColor: '#0F172A', borderColor: '#0EA5E9', color: '#F1F5F9' }}
                  />
                </div>
              </div>

              {/* Team Information */}
              <div className="p-6 rounded-lg" style={{ backgroundColor: '#1E293B' }}>
                <h3 className="text-lg font-bold mb-4" style={{ color: '#F1F5F9' }}>Team Information</h3>
                <div className="space-y-4">
                  <div>
                    <label className="block text-sm mb-2" style={{ color: '#CBD5E1' }}>Number of Employees</label>
                    <input
                      type="number"
                      value={employeeCount}
                      onChange={handleEmployeeCountChange}
                      min="1"
                      className="w-full px-4 py-3 rounded-lg border-2"
                      style={{ backgroundColor: '#0F172A', borderColor: '#0EA5E9', color: '#F1F5F9' }}
                    />
                  </div>

                  <div>
                    <label className="block text-sm mb-2" style={{ color: '#CBD5E1' }}>Salary Input Method</label>
                    <div className="flex gap-4">
                      <label className="flex items-center gap-2 cursor-pointer">
                        <input
                          type="radio"
                          value="average"
                          checked={salaryType === 'average'}
                          onChange={(e) => setSalaryType(e.target.value)}
                        />
                        <span style={{ color: '#F1F5F9' }} className="text-sm">Average</span>
                      </label>
                      <label className="flex items-center gap-2 cursor-pointer">
                        <input
                          type="radio"
                          value="individual"
                          checked={salaryType === 'individual'}
                          onChange={(e) => setSalaryType(e.target.value)}
                        />
                        <span style={{ color: '#F1F5F9' }} className="text-sm">Individual</span>
                      </label>
                    </div>
                  </div>

                  {salaryType === 'average' ? (
                    <div>
                      <label className="block text-sm mb-2" style={{ color: '#CBD5E1' }}>Average Annual Salary ($)</label>
                      <input
                        type="number"
                        value={averageSalary}
                        onChange={(e) => setAverageSalary(parseFloat(e.target.value) || 0)}
                        className="w-full px-4 py-3 rounded-lg border-2"
                        style={{ backgroundColor: '#0F172A', borderColor: '#0EA5E9', color: '#F1F5F9' }}
                      />
                    </div>
                  ) : (
                    <div className="space-y-2">
                      {employees.map((emp, index) => (
                        <div key={index}>
                          <label className="block text-xs mb-1" style={{ color: '#CBD5E1' }}>Employee {index + 1} ($)</label>
                          <input
                            type="number"
                            value={emp.salary}
                            onChange={(e) => handleEmployeeSalaryChange(index, e.target.value)}
                            className="w-full px-3 py-2 rounded-lg border-2 text-sm"
                            style={{ backgroundColor: '#0F172A', borderColor: '#0EA5E9', color: '#F1F5F9' }}
                          />
                        </div>
                      ))}
                    </div>
                  )}
                </div>
              </div>

              {/* Activities */}
              <div className="p-6 rounded-lg" style={{ backgroundColor: '#1E293B' }}>
                <h3 className="text-lg font-bold mb-4" style={{ color: '#F1F5F9' }}>Hours Saved Per Activity</h3>
                <div className="space-y-3">
                  {activities.map((activity, index) => (
                    <div key={index} className="flex gap-2 items-end">
                      <div className="flex-1">
                        <label className="block text-xs mb-1" style={{ color: '#CBD5E1' }}>Name</label>
                        <input
                          type="text"
                          value={activity.name}
                          onChange={(e) => handleActivityChange(index, 'name', e.target.value)}
                          placeholder="Activity"
                          className="w-full px-3 py-2 rounded-lg border-2 text-sm"
                          style={{ backgroundColor: '#0F172A', borderColor: '#0EA5E9', color: '#F1F5F9' }}
                        />
                      </div>
                      <div className="w-24">
                        <label className="block text-xs mb-1" style={{ color: '#CBD5E1' }}>Hours/Day</label>
                        <input
                          type="number"
                          value={activity.hoursSavedPerDay}
                          onChange={(e) => handleActivityChange(index, 'hoursSavedPerDay', e.target.value)}
                          step="0.5"
                          className="w-full px-3 py-2 rounded-lg border-2 text-sm"
                          style={{ backgroundColor: '#0F172A', borderColor: '#0EA5E9', color: '#F1F5F9' }}
                        />
                      </div>
                      {activities.length > 1 && (
                        <button
                          onClick={() => removeActivity(index)}
                          className="px-3 py-2 rounded-lg text-sm font-medium"
                          style={{ backgroundColor: '#0C4F64', color: '#FCD34D' }}
                        >
                          ×
                        </button>
                      )}
                    </div>
                  ))}
                  <button
                    onClick={addActivity}
                    className="w-full mt-3 px-4 py-2 rounded-lg font-medium text-sm transition"
                    style={{ backgroundColor: '#0EA5E9', color: '#F1F5F9' }}
                  >
                    + Add Activity
                  </button>
                </div>
              </div>
            </div>

            {/* RIGHT SIDE - RESULTS */}
            <div className="space-y-6">
              {/* Key Metrics */}
              <div className="grid grid-cols-2 gap-4">
                <div className="p-6 rounded-lg border" style={{ backgroundColor: '#1E293B', borderColor: '#0EA5E9' }}>
                  <div className="flex items-center gap-2 mb-2">
                    <DollarSign size={18} style={{ color: '#06B6D4' }} />
                    <p style={{ color: '#CBD5E1' }} className="text-sm">Annual Benefit</p>
                  </div>
                  <p className="text-2xl font-bold" style={{ color: '#06B6D4' }}>
                    ${totalBenefit.toLocaleString('en-US', { maximumFractionDigits: 0 })}
                  </p>
                </div>

                <div className="p-6 rounded-lg border" style={{ backgroundColor: '#1E293B', borderColor: '#0EA5E9' }}>
                  <div className="flex items-center gap-2 mb-2">
                    <TrendingUp size={18} style={{ color: '#06B6D4' }} />
                    <p style={{ color: '#CBD5E1' }} className="text-sm">ROI</p>
                  </div>
                  <p className="text-2xl font-bold" style={{ color: '#FCD34D' }}>
                    {roi}%
                  </p>
                </div>

                <div className="p-6 rounded-lg border" style={{ backgroundColor: '#1E293B', borderColor: '#0EA5E9' }}>
                  <div className="flex items-center gap-2 mb-2">
                    <Clock size={18} style={{ color: '#06B6D4' }} />
                    <p style={{ color: '#CBD5E1' }} className="text-sm">Break-Even</p>
                  </div>
                  <p className="text-2xl font-bold" style={{ color: '#06B6D4' }}>
                    {breakEvenDays} days
                  </p>
                </div>

                <div className="p-6 rounded-lg border" style={{ backgroundColor: '#1E293B', borderColor: '#0EA5E9' }}>
                  <div className="flex items-center gap-2 mb-2">
                    <DollarSign size={18} style={{ color: '#06B6D4' }} />
                    <p style={{ color: '#CBD5E1' }} className="text-sm">Net Benefit (Y1)</p>
                  </div>
                  <p className="text-2xl font-bold" style={{ color: '#FCD34D' }}>
                    ${netBenefit.toLocaleString('en-US', { maximumFractionDigits: 0 })}
                  </p>
                </div>
              </div>

              {/* Benefit Breakdown */}
              <div className="p-6 rounded-lg" style={{ backgroundColor: '#1E293B', borderLeft: '4px solid #06B6D4' }}>
                <h3 className="text-lg font-bold mb-4" style={{ color: '#F1F5F9' }}>Benefit Breakdown</h3>
                <div className="space-y-3">
                  <div className="flex justify-between items-center">
                    <span style={{ color: '#CBD5E1' }} className="text-sm">Hours Saved Per Year</span>
                    <span style={{ color: '#06B6D4' }} className="font-semibold text-sm">
                      {totalHoursSaved.toLocaleString('en-US', { maximumFractionDigits: 0 })} hrs
                    </span>
                  </div>
                  <div className="flex justify-between items-center">
                    <span style={{ color: '#CBD5E1' }} className="text-sm">Average Hourly Rate</span>
                    <span style={{ color: '#06B6D4' }} className="font-semibold text-sm">
                      ${averageHourlyRate.toFixed(2)}/hr
                    </span>
                  </div>
                  <div className="flex justify-between items-center">
                    <span style={{ color: '#CBD5E1' }} className="text-sm">Cost Per Hour Saved</span>
                    <span style={{ color: '#06B6D4' }} className="font-semibold text-sm">
                      ${costPerHour.toFixed(2)}/hr
                    </span>
                  </div>
                  <div className="flex justify-between items-center">
                    <span style={{ color: '#CBD5E1' }} className="text-sm">Monthly Benefit</span>
                    <span style={{ color: '#06B6D4' }} className="font-semibold text-sm">
                      ${monthlyBenefit.toLocaleString('en-US', { maximumFractionDigits: 0 })}
                    </span>
                  </div>
                  <div className="border-t pt-3 mt-3" style={{ borderColor: '#0C4F64' }}>
                    <div className="flex justify-between items-center">
                      <span style={{ color: '#F1F5F9' }} className="font-semibold text-sm">Total Annual Benefit</span>
                      <span style={{ color: '#FCD34D' }} className="text-lg font-bold">
                        ${totalBenefit.toLocaleString('en-US', { maximumFractionDigits: 0 })}
                      </span>
                    </div>
                  </div>
                </div>
              </div>

              {/* Key Insight */}
              <div className="p-6 rounded-lg border-2" style={{ backgroundColor: '#0C4F64', borderColor: '#06B6D4' }}>
                <div className="flex gap-3">
                  <AlertCircle size={20} style={{ color: '#06B6D4', flexShrink: 0 }} />
                  <div>
                    <p style={{ color: '#F1F5F9' }} className="font-semibold text-sm mb-1">Key Insight</p>
                    <p style={{ color: '#CBD5E1' }} className="text-sm">
                      For every $1 invested, you get ${(totalBenefit / trainingCost).toFixed(2)} in return. Your investment pays for itself in {breakEvenDays} days.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        )}

        {/* BREAK-EVEN TAB */}
        {activeTab === 'breakeven' && (
          <div className="space-y-8">
            <div className="grid grid-cols-3 gap-4">
              <div className="p-6 rounded-lg" style={{ backgroundColor: '#1E293B', borderLeft: '4px solid #06B6D4' }}>
                <p style={{ color: '#CBD5E1' }} className="text-sm mb-2">Investment</p>
                <p className="text-3xl font-bold" style={{ color: '#F1F5F9' }}>
                  ${trainingCost.toLocaleString('en-US', { maximumFractionDigits: 0 })}
                </p>
              </div>
              <div className="p-6 rounded-lg" style={{ backgroundColor: '#1E293B', borderLeft: '4px solid #06B6D4' }}>
                <p style={{ color: '#CBD5E1' }} className="text-sm mb-2">Monthly Benefit</p>
                <p className="text-3xl font-bold" style={{ color: '#06B6D4' }}>
                  ${monthlyBenefit.toLocaleString('en-US', { maximumFractionDigits: 0 })}
                </p>
              </div>
              <div className="p-6 rounded-lg" style={{ backgroundColor: '#1E293B', borderLeft: '4px solid #FCD34D' }}>
                <p style={{ color: '#CBD5E1' }} className="text-sm mb-2">Break-Even</p>
                <p className="text-3xl font-bold" style={{ color: '#FCD34D' }}>
                  {breakEvenDays} days
                </p>
              </div>
            </div>

            <div className="p-8 rounded-lg" style={{ backgroundColor: '#1E293B' }}>
              <h3 className="text-lg font-bold mb-6" style={{ color: '#F1F5F9' }}>Cumulative Benefit Timeline</h3>
              <BreakEvenTimeline />
            </div>

            <div className="p-8 rounded-lg" style={{ backgroundColor: '#0C4F64' }}>
              <h3 className="text-lg font-bold mb-4" style={{ color: '#06B6D4' }}>What This Means</h3>
              <ul className="space-y-3" style={{ color: '#CBD5E1' }}>
                <li className="text-sm">✓ Investment fully recouped in {breakEvenDays} days</li>
                <li className="text-sm">✓ Month 1: ${(monthlyBenefit - trainingCost).toLocaleString('en-US', { maximumFractionDigits: 0 })} net profit</li>
                <li className="text-sm">✓ Year 1: ${netBenefit.toLocaleString('en-US', { maximumFractionDigits: 0 })} total benefit</li>
                <li className="text-sm">✓ Year-over-year: Unlimited benefit with no additional training cost</li>
              </ul>
            </div>
          </div>
        )}
      </div>

      {/* Footer */}
      <div className="border-t py-8 mt-16" style={{ borderColor: '#1E293B', backgroundColor: '#0F172A' }}>
        <div className="max-w-7xl mx-auto px-6">
          <div className="grid grid-cols-2 gap-8 mb-8">
            {/* Left: About */}
            <div style={{ color: '#CBD5E1' }}>
              <p className="text-sm mb-2">Calculator based on Wayne Cascio's Investing in People Framework</p>
              <p className="text-xs">Annual work days: 250 | Assumes 2,080 hours per year (52 weeks × 40 hours)</p>
            </div>

            {/* Right: Contact */}
            <div className="text-right">
              <p className="text-sm font-semibold mb-3" style={{ color: '#FCD34D' }}>Designed by Violetta Drobot</p>
              <div className="flex gap-4 justify-end">
                <a
                  href="https://www.linkedin.com/in/violetta-drobot-ms-in-hrm-and-pm-shrm-scp/"
                  target="_blank"
                  rel="noopener noreferrer"
                  className="flex items-center gap-2 hover:opacity-80 transition"
                  style={{ color: '#06B6D4' }}
                >
                  <Linkedin size={18} />
                  <span className="text-sm">LinkedIn</span>
                </a>
                <a
                  href="mailto:violettadrobot@gmail.com"
                  className="flex items-center gap-2 hover:opacity-80 transition"
                  style={{ color: '#06B6D4' }}
                >
                  <Mail size={18} />
                  <span className="text-sm">Email</span>
                </a>
              </div>
            </div>
          </div>

          {/* Copyright */}
          <div className="border-t pt-6 text-center" style={{ borderColor: '#1E293B', color: '#CBD5E1' }}>
            <p className="text-xs">© Violetta Drobot - AI Compliance Consultant</p>
          </div>
        </div>
      </div>
    </div>
  );
}
