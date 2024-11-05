import React, { useState, useEffect } from 'react';

const MathMatchingGame = () => {
  const [difficulty, setDifficulty] = useState('קל');
  const [exercises, setExercises] = useState([]);
  const [selectedExercise, setSelectedExercise] = useState(null);
  const [showSuccess, setShowSuccess] = useState(false);
  const [showError, setShowError] = useState(false);
  const [matchedPairs, setMatchedPairs] = useState([]);

  const generateExercises = (difficulty) => {
    let range, numPairs;
    
    switch(difficulty) {
      case 'קל':
        range = { min: 1, max: 10 };
        numPairs = 4;
        break;
      case 'בינוני':
        range = { min: 10, max: 50 };
        numPairs = 6;
        break;
      case 'קשה':
        range = { min: 50, max: 100 };
        numPairs = 8;
        break;
      default:
        range = { min: 1, max: 10 };
        numPairs = 4;
    }

    const pairs = [];
    for (let i = 0; i < numPairs; i++) {
      const num1 = Math.floor(Math.random() * (range.max - range.min + 1)) + range.min;
      const num2 = Math.floor(Math.random() * (range.max - range.min + 1)) + range.min;
      const result = num1 + num2;
      pairs.push({
        id: i,
        exercise: `${num1} + ${num2}`,
        result: result.toString()
      });
    }

    const flatExercises = pairs.flatMap(pair => [
      { id: `ex-${pair.id}`, value: pair.exercise, pairId: pair.id, type: 'exercise' },
      { id: `res-${pair.id}`, value: pair.result, pairId: pair.id, type: 'result' }
    ]);

    return flatExercises.sort(() => Math.random() - 0.5);
  };

  useEffect(() => {
    setExercises(generateExercises(difficulty));
    setMatchedPairs([]);
    setSelectedExercise(null);
  }, [difficulty]);

  const handleExerciseClick = (exercise) => {
    if (matchedPairs.includes(exercise.pairId)) return;
    
    if (!selectedExercise) {
      setSelectedExercise(exercise);
    } else {
      if (selectedExercise.id === exercise.id) return;
      
      if (selectedExercise.pairId === exercise.pairId) {
        setMatchedPairs([...matchedPairs, exercise.pairId]);
        setShowSuccess(true);
        setTimeout(() => setShowSuccess(false), 1000);
      } else {
        setShowError(true);
        setTimeout(() => setShowError(false), 1000);
      }
      setSelectedExercise(null);
    }
  };

  // חישוב מספר העמודות בהתאם לרמת הקושי
  const getGridColumns = () => {
    switch(difficulty) {
      case 'קל': return 'grid-cols-2 sm:grid-cols-4';
      case 'בינוני': return 'grid-cols-2 sm:grid-cols-3 md:grid-cols-4';
      case 'קשה': return 'grid-cols-2 sm:grid-cols-3 md:grid-cols-4';
      default: return 'grid-cols-2 sm:grid-cols-4';
    }
  };

  return (
    <div className="p-2 sm:p-4 max-w-4xl mx-auto">
      {/* כפתורי רמת קושי */}
      <div className="flex flex-wrap gap-2 mb-4 justify-center">
        {['קל', 'בינוני', 'קשה'].map((level) => (
          <button
            key={level}
            onClick={() => setDifficulty(level)}
            className={`px-3 py-2 text-sm sm:text-base sm:px-4 sm:py-2 rounded-lg ${
              difficulty === level
                ? 'bg-blue-500 text-white'
                : 'bg-gray-200 hover:bg-gray-300'
            } touch-manipulation`}
          >
            {level}
          </button>
        ))}
      </div>

      {/* רשת התרגילים */}
      <div className={`grid ${getGridColumns()} gap-2 sm:gap-4`}>
        {exercises.map((exercise) => (
          <button
            key={exercise.id}
            onClick={() => handleExerciseClick(exercise)}
            className={`p-3 sm:p-4 text-base sm:text-lg rounded-lg transition-all 
              ${matchedPairs.includes(exercise.pairId)
                ? 'bg-green-200 cursor-default'
                : selectedExercise?.id === exercise.id
                ? 'bg-blue-200'
                : 'bg-white hover:bg-gray-100'
              } border-2 border-gray-300 min-h-[3rem] sm:min-h-[4rem] 
              touch-manipulation active:scale-95`}
            disabled={matchedPairs.includes(exercise.pairId)}
          >
            {exercise.value}
          </button>
        ))}
      </div>

      {/* הודעות משוב */}
      <div className="fixed bottom-4 right-4 left-4 flex justify-center">
        {showSuccess && (
          <div className="bg-green-500 text-white px-4 py-2 rounded-lg shadow text-center w-full max-w-xs">
            תשובה נכונה!
          </div>
        )}

        {showError && (
          <div className="bg-red-500 text-white px-4 py-2 rounded-lg shadow text-center w-full max-w-xs">
            טעות! נסה שוב
          </div>
        )}
      </div>
    </div>
  );
};

export default MathMatchingGame;
