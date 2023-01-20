# nge-to-left


stack<int> st;
	
	ngl[0] = -1;
	st.push(a[0]);
	for (int i = 1; i < n; i++) {
		while (st.size() > 0 && a[i] > st.top()) {
			st.pop();
		}
		if (st.size() == 0) {
			ngl[i] = -1;
		}
		else {
			ngl[i] = st.top();
		}
		st.push(a[i]);
	}
	while (st.size() > 0) {
		st.pop();
	}

	
